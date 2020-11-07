---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890122"
---
# <span data-ttu-id="7d9b5-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7d9b5-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="7d9b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9b5-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="7d9b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d9b5-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d9b5-105">DESCRIPTION</span></span>
<span data-ttu-id="7d9b5-106">Polecenie cmdlet **Add-AzVMAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="7d9b5-107">Określ dodatkowe kodowanie Base 64 informacje o formacie XML, które to polecenie cmdlet dodaje do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="7d9b5-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d9b5-108">EXAMPLES</span></span>

### <span data-ttu-id="7d9b5-109">Przykład 1: dodawanie zawartości do unattend.xml</span><span class="sxs-lookup"><span data-stu-id="7d9b5-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="7d9b5-110">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="7d9b5-111">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7d9b5-112">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="7d9b5-113">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="7d9b5-114">Trzecie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="7d9b5-115">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="7d9b5-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="7d9b5-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="7d9b5-117">W czwartym poleceniu użyto polecenia cmdlet **Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7d9b5-118">W piątym poleceniu jest przypisywana zawartość zmiennej $AucContent.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="7d9b5-119">Zawartość zawiera hasło.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-119">The content includes a password.</span></span>

<span data-ttu-id="7d9b5-120">Polecenie ostatnie powoduje dodanie zawartości przechowywanej w $AucContent do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="7d9b5-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d9b5-121">PARAMETERS</span></span>

### <span data-ttu-id="7d9b5-122">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="7d9b5-122">-Content</span></span>
<span data-ttu-id="7d9b5-123">Określa zakodowaną w podstawie 64 zawartość w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="7d9b5-124">To polecenie cmdlet umożliwia dodanie zawartości do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="7d9b5-125">Zawartość XML musi być mniejsza niż 4 KB i musi zawierać element główny ustawienia lub funkcję, które zostaną wstawione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="7d9b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9b5-126">-DefaultProfile</span></span>
<span data-ttu-id="7d9b5-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9b5-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="7d9b5-128">-SettingName</span></span>
<span data-ttu-id="7d9b5-129">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="7d9b5-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7d9b5-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d9b5-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="7d9b5-131">FirstLogonCommands</span></span>
- <span data-ttu-id="7d9b5-132">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="7d9b5-132">AutoLogon</span></span>

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

### <span data-ttu-id="7d9b5-133">-VM</span><span class="sxs-lookup"><span data-stu-id="7d9b5-133">-VM</span></span>
<span data-ttu-id="7d9b5-134">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="7d9b5-135">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9b5-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="7d9b5-136">Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7d9b5-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="7d9b5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9b5-137">CommonParameters</span></span>
<span data-ttu-id="7d9b5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9b5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9b5-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9b5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9b5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d9b5-140">INPUTS</span></span>

### <span data-ttu-id="7d9b5-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7d9b5-141">PSVirtualMachine</span></span>
<span data-ttu-id="7d9b5-142">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="7d9b5-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7d9b5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d9b5-143">OUTPUTS</span></span>

### <span data-ttu-id="7d9b5-144">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7d9b5-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7d9b5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d9b5-145">NOTES</span></span>

## <span data-ttu-id="7d9b5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d9b5-146">RELATED LINKS</span></span>

[<span data-ttu-id="7d9b5-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="7d9b5-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="7d9b5-148">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7d9b5-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7d9b5-149">Nowe — AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7d9b5-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
