---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238990"
---
# <span data-ttu-id="d971f-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d971f-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="d971f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d971f-102">SYNOPSIS</span></span>
<span data-ttu-id="d971f-103">Umożliwia dodanie informacji do nienadzorowanych plików odpowiedzi Instalatora systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d971f-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d971f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d971f-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d971f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d971f-105">DESCRIPTION</span></span>
<span data-ttu-id="d971f-106">Polecenie **cmdlet Add-AzVMAdditionalUnattendContent** umożliwia dodanie informacji do nienadzorowanych plików odpowiedzi Instalatora systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="d971f-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="d971f-107">Określ dodatkowe informacje w formacie xml z kodem base 64, które to polecenie cmdlet dodaje do unattend.xml pliku.</span><span class="sxs-lookup"><span data-stu-id="d971f-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="d971f-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d971f-108">EXAMPLES</span></span>

### <span data-ttu-id="d971f-109">Przykład 1. Dodawanie zawartości do unattend.xml</span><span class="sxs-lookup"><span data-stu-id="d971f-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="d971f-110">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.</span><span class="sxs-lookup"><span data-stu-id="d971f-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="d971f-111">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.</span><span class="sxs-lookup"><span data-stu-id="d971f-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d971f-112">To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d971f-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d971f-113">Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d971f-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="d971f-114">Trzecie polecenie tworzy obiekt poświadczeń za pomocą Get-Credential cmdlet, a następnie zapisuje wynik w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="d971f-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="d971f-115">Polecenie monituje o nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="d971f-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="d971f-116">Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d971f-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="d971f-117">Czwarte polecenie używa polecenia **cmdlet Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d971f-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d971f-118">Piąte polecenie przypisuje zawartość do zmiennej $AucContent danych.</span><span class="sxs-lookup"><span data-stu-id="d971f-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="d971f-119">Zawartość zawiera hasło.</span><span class="sxs-lookup"><span data-stu-id="d971f-119">The content includes a password.</span></span>
<span data-ttu-id="d971f-120">Ostatnie polecenie dodaje zawartość przechowywaną w pliku $AucContent do unattend.xml pliku.</span><span class="sxs-lookup"><span data-stu-id="d971f-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="d971f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d971f-121">PARAMETERS</span></span>

### <span data-ttu-id="d971f-122">— Zawartość</span><span class="sxs-lookup"><span data-stu-id="d971f-122">-Content</span></span>
<span data-ttu-id="d971f-123">Określa zawartość zakodowaną w formacie XML o podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="d971f-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="d971f-124">To polecenie cmdlet dodaje zawartość do unattend.xml pliku.</span><span class="sxs-lookup"><span data-stu-id="d971f-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="d971f-125">Zawartość XML musi mieć mniej niż 4 KB i musi zawierać element główny ustawienia lub funkcji wstawianych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d971f-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d971f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d971f-126">-DefaultProfile</span></span>
<span data-ttu-id="d971f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d971f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d971f-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d971f-128">-SettingName</span></span>
<span data-ttu-id="d971f-129">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="d971f-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d971f-130">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d971f-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d971f-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d971f-131">FirstLogonCommands</span></span>
- <span data-ttu-id="d971f-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="d971f-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d971f-133">- MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="d971f-133">-VM</span></span>
<span data-ttu-id="d971f-134">Określa obiekt maszyny wirtualnej, który zostanie zmodyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d971f-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d971f-135">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="d971f-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d971f-136">Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="d971f-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d971f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d971f-137">CommonParameters</span></span>
<span data-ttu-id="d971f-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d971f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d971f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d971f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d971f-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d971f-140">INPUTS</span></span>

### <span data-ttu-id="d971f-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d971f-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d971f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d971f-142">System.String</span></span>

### <span data-ttu-id="d971f-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d971f-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d971f-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d971f-144">OUTPUTS</span></span>

### <span data-ttu-id="d971f-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d971f-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d971f-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d971f-146">NOTES</span></span>

## <span data-ttu-id="d971f-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d971f-147">RELATED LINKS</span></span>

[<span data-ttu-id="d971f-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d971f-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d971f-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d971f-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d971f-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d971f-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
