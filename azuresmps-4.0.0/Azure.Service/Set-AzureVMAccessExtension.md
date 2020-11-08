---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054777"
---
# <span data-ttu-id="8e940-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8e940-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="8e940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e940-102">SYNOPSIS</span></span>
<span data-ttu-id="8e940-103">Ustawia rozszerzenie VMAccess dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="8e940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e940-104">SYNTAX</span></span>

### <span data-ttu-id="8e940-105">EnableAccessExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e940-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e940-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8e940-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8e940-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8e940-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8e940-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e940-108">DESCRIPTION</span></span>
<span data-ttu-id="8e940-109">Polecenie cmdlet **Set-AzureVMAccessExtension** dodaje rozszerzenie VMAccess maszyny wirtualnej do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="8e940-110">Za pomocą rozszerzenia VMAccess można ustawić hasło tymczasowe i należy je natychmiast zmienić po zalogowaniu się do komputera.</span><span class="sxs-lookup"><span data-stu-id="8e940-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="8e940-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e940-111">EXAMPLES</span></span>

### <span data-ttu-id="8e940-112">Przykład 1: Ustawianie rozszerzenia VMAccess zastosowanego do określonej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8e940-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="8e940-113">To polecenie ustawia rozszerzenie VMAccess zastosowane do określonej maszyny wirtualnej jako przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="8e940-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="8e940-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e940-114">PARAMETERS</span></span>

### <span data-ttu-id="8e940-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="8e940-115">-Disable</span></span>
<span data-ttu-id="8e940-116">Wskazuje, że to polecenie cmdlet powoduje wyłączenie stanu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8e940-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="8e940-117">-ForceUpdate</span></span>
<span data-ttu-id="8e940-118">Wskazuje, że ten aplet polecenia ponownie zastosuje konfigurację do rozszerzenia, gdy konfiguracja nie została zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="8e940-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8e940-119">-InformationAction</span></span>
<span data-ttu-id="8e940-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="8e940-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8e940-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8e940-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e940-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="8e940-122">Continue</span></span>
- <span data-ttu-id="8e940-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="8e940-123">Ignore</span></span>
- <span data-ttu-id="8e940-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="8e940-124">Inquire</span></span>
- <span data-ttu-id="8e940-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8e940-125">SilentlyContinue</span></span>
- <span data-ttu-id="8e940-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="8e940-126">Stop</span></span>
- <span data-ttu-id="8e940-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="8e940-127">Suspend</span></span>

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

### <span data-ttu-id="8e940-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8e940-128">-InformationVariable</span></span>
<span data-ttu-id="8e940-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="8e940-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8e940-130">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="8e940-130">-Password</span></span>
<span data-ttu-id="8e940-131">Określa hasło do resetowania poświadczeń maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="8e940-132">-Profile</span></span>
<span data-ttu-id="8e940-133">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e940-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e940-134">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8e940-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e940-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="8e940-135">-ReferenceName</span></span>
<span data-ttu-id="8e940-136">Określa nazwę referencyjną rozszerzenia programu Access.</span><span class="sxs-lookup"><span data-stu-id="8e940-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="8e940-137">Jest to ciąg zdefiniowany przez użytkownika, który służy do odwoływania się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8e940-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="8e940-138">Jest ona określana po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="8e940-139">W przypadku kolejnych aktualizacji należy określić poprzednio zastosowaną nazwę referencyjną podczas aktualizowania rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8e940-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="8e940-140">Element *ReferenceName* przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="8e940-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-141">— Odinstalowywanie</span><span class="sxs-lookup"><span data-stu-id="8e940-141">-Uninstall</span></span>
<span data-ttu-id="8e940-142">Wskazuje, czy to polecenie cmdlet Odinstalowuje rozszerzenie programu Access.</span><span class="sxs-lookup"><span data-stu-id="8e940-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="8e940-143">-UserName</span></span>
<span data-ttu-id="8e940-144">Określa nazwę użytkownika, za pomocą którego to polecenie cmdlet resetuje poświadczenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-145">-Version</span><span class="sxs-lookup"><span data-stu-id="8e940-145">-Version</span></span>
<span data-ttu-id="8e940-146">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="8e940-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e940-147">-VM</span><span class="sxs-lookup"><span data-stu-id="8e940-147">-VM</span></span>
<span data-ttu-id="8e940-148">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8e940-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="8e940-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e940-149">CommonParameters</span></span>
<span data-ttu-id="8e940-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e940-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e940-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e940-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e940-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e940-152">INPUTS</span></span>

## <span data-ttu-id="8e940-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e940-153">OUTPUTS</span></span>

## <span data-ttu-id="8e940-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e940-154">NOTES</span></span>

## <span data-ttu-id="8e940-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e940-155">RELATED LINKS</span></span>

[<span data-ttu-id="8e940-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8e940-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="8e940-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8e940-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


