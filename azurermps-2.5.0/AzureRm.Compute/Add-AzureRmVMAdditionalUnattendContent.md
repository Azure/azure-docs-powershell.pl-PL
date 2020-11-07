---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmadditionalunattendcontent
schema: 2.0.0
ms.openlocfilehash: e1441178898f675d0ccc5e654d3020212e532d90
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899005"
---
# <span data-ttu-id="c8914-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="c8914-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="c8914-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8914-102">SYNOPSIS</span></span>
<span data-ttu-id="c8914-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c8914-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8914-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8914-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8914-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c8914-105">DESCRIPTION</span></span>
<span data-ttu-id="c8914-106">Polecenie cmdlet **Add-AzureRmVMAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="c8914-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="c8914-107">Określ dodatkowe kodowanie Base 64 informacje o formacie XML, które to polecenie cmdlet dodaje do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="c8914-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="c8914-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8914-108">EXAMPLES</span></span>

### <span data-ttu-id="c8914-109">Przykład 1: dodawanie zawartości do unattend.xml</span><span class="sxs-lookup"><span data-stu-id="c8914-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="c8914-110">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c8914-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="c8914-111">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c8914-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c8914-112">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c8914-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c8914-113">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="c8914-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="c8914-114">Trzecie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="c8914-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="c8914-115">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="c8914-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="c8914-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="c8914-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="c8914-117">W czwartym poleceniu użyto polecenia cmdlet **Set-AzureRmVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c8914-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="c8914-118">W piątym poleceniu jest przypisywana zawartość zmiennej $AucContent.</span><span class="sxs-lookup"><span data-stu-id="c8914-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="c8914-119">Zawartość zawiera hasło.</span><span class="sxs-lookup"><span data-stu-id="c8914-119">The content includes a password.</span></span>

<span data-ttu-id="c8914-120">Polecenie ostatnie powoduje dodanie zawartości przechowywanej w $AucContent do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="c8914-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="c8914-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8914-121">PARAMETERS</span></span>

### <span data-ttu-id="c8914-122">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="c8914-122">-Content</span></span>
<span data-ttu-id="c8914-123">Określa zakodowaną w podstawie 64 zawartość w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="c8914-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="c8914-124">To polecenie cmdlet umożliwia dodanie zawartości do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="c8914-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="c8914-125">Zawartość XML musi być mniejsza niż 4 KB i musi zawierać element główny ustawienia lub funkcję, które zostaną wstawione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8914-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="c8914-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8914-126">-DefaultProfile</span></span>
<span data-ttu-id="c8914-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8914-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8914-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="c8914-128">-SettingName</span></span>
<span data-ttu-id="c8914-129">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="c8914-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="c8914-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c8914-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8914-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="c8914-131">FirstLogonCommands</span></span>
- <span data-ttu-id="c8914-132">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="c8914-132">AutoLogon</span></span>

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

### <span data-ttu-id="c8914-133">-VM</span><span class="sxs-lookup"><span data-stu-id="c8914-133">-VM</span></span>
<span data-ttu-id="c8914-134">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8914-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="c8914-135">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="c8914-135">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="c8914-136">Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="c8914-136">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="c8914-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8914-137">CommonParameters</span></span>
<span data-ttu-id="c8914-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8914-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8914-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8914-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8914-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8914-140">INPUTS</span></span>

### <span data-ttu-id="c8914-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8914-141">PSVirtualMachine</span></span>
<span data-ttu-id="c8914-142">Parametr "VM" akceptuje wartość typu "PSVirtualMachine" z procesu</span><span class="sxs-lookup"><span data-stu-id="c8914-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c8914-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8914-143">OUTPUTS</span></span>

### <span data-ttu-id="c8914-144">Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c8914-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c8914-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8914-145">NOTES</span></span>

## <span data-ttu-id="c8914-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8914-146">RELATED LINKS</span></span>

[<span data-ttu-id="c8914-147">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c8914-147">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="c8914-148">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c8914-148">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="c8914-149">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c8914-149">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
