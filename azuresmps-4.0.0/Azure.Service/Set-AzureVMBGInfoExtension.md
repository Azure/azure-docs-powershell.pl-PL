---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055009"
---
# <span data-ttu-id="34244-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="34244-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="34244-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34244-102">SYNOPSIS</span></span>
<span data-ttu-id="34244-103">Ustawia rozszerzenie BGInfo dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34244-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="34244-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34244-104">SYNTAX</span></span>

### <span data-ttu-id="34244-105">SetBGInfoExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34244-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="34244-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="34244-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="34244-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34244-107">DESCRIPTION</span></span>
<span data-ttu-id="34244-108">Polecenie cmdlet **Set-AzureVMBGInfoExtension** ustawia rozszerzenie BgInfo maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34244-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="34244-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34244-109">EXAMPLES</span></span>

### <span data-ttu-id="34244-110">Przykład 1: Ustawianie rozszerzenia BGInfo dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="34244-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="34244-111">To polecenie ustawia rozszerzenie BGInfo dla określonej maszyny wirtualnej jako przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="34244-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="34244-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34244-112">PARAMETERS</span></span>

### <span data-ttu-id="34244-113">-Disable</span><span class="sxs-lookup"><span data-stu-id="34244-113">-Disable</span></span>
<span data-ttu-id="34244-114">Wskazuje, że to polecenie cmdlet wyłącza stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="34244-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34244-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="34244-115">-InformationAction</span></span>
<span data-ttu-id="34244-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="34244-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="34244-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="34244-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34244-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="34244-118">Continue</span></span>
- <span data-ttu-id="34244-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="34244-119">Ignore</span></span>
- <span data-ttu-id="34244-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="34244-120">Inquire</span></span>
- <span data-ttu-id="34244-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="34244-121">SilentlyContinue</span></span>
- <span data-ttu-id="34244-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="34244-122">Stop</span></span>
- <span data-ttu-id="34244-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="34244-123">Suspend</span></span>

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

### <span data-ttu-id="34244-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="34244-124">-InformationVariable</span></span>
<span data-ttu-id="34244-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="34244-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="34244-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="34244-126">-Profile</span></span>
<span data-ttu-id="34244-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34244-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34244-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="34244-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34244-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="34244-129">-ReferenceName</span></span>
<span data-ttu-id="34244-130">Określa nazwę referencyjną rozszerzenia BGInfo.</span><span class="sxs-lookup"><span data-stu-id="34244-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="34244-131">Ten parametr jest ciągiem zdefiniowanym przez użytkownika, którego można używać w celu odwoływania się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="34244-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="34244-132">Jest ona określana po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34244-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="34244-133">Podczas aktualizowania rozszerzenia możesz określić poprzednio zastosowaną nazwę referencyjną.</span><span class="sxs-lookup"><span data-stu-id="34244-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34244-134">— Odinstalowywanie</span><span class="sxs-lookup"><span data-stu-id="34244-134">-Uninstall</span></span>
<span data-ttu-id="34244-135">Wskazuje, że to polecenie cmdlet Odinstalowuje rozszerzenie BGInfo.</span><span class="sxs-lookup"><span data-stu-id="34244-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34244-136">-Version</span><span class="sxs-lookup"><span data-stu-id="34244-136">-Version</span></span>
<span data-ttu-id="34244-137">Określa wersję rozszerzenia BGInfo.</span><span class="sxs-lookup"><span data-stu-id="34244-137">Specifies the version of the BGInfo extension.</span></span>

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

### <span data-ttu-id="34244-138">-VM</span><span class="sxs-lookup"><span data-stu-id="34244-138">-VM</span></span>
<span data-ttu-id="34244-139">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34244-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="34244-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34244-140">CommonParameters</span></span>
<span data-ttu-id="34244-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34244-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34244-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34244-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34244-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34244-143">INPUTS</span></span>

## <span data-ttu-id="34244-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34244-144">OUTPUTS</span></span>

## <span data-ttu-id="34244-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34244-145">NOTES</span></span>

## <span data-ttu-id="34244-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34244-146">RELATED LINKS</span></span>

[<span data-ttu-id="34244-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="34244-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="34244-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="34244-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


