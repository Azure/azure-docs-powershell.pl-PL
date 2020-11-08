---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054815"
---
# <span data-ttu-id="b17f5-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="b17f5-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="b17f5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b17f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b17f5-103">Ustawia rozszerzenie Puppet dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b17f5-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="b17f5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b17f5-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b17f5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b17f5-105">DESCRIPTION</span></span>
<span data-ttu-id="b17f5-106">Polecenie cmdlet **Set-AzureVMPuppetExtension** ustawia rozszerzenie Puppet maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b17f5-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="b17f5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b17f5-107">EXAMPLES</span></span>

### <span data-ttu-id="b17f5-108">Przykład 1: Ustawianie rozszerzenia Puppet dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="b17f5-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="b17f5-109">W tym przykładzie ustawiono rozszerzenie Puppet dla określonej maszyny wirtualnej jako przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="b17f5-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="b17f5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b17f5-110">PARAMETERS</span></span>

### <span data-ttu-id="b17f5-111">-Disable</span><span class="sxs-lookup"><span data-stu-id="b17f5-111">-Disable</span></span>
<span data-ttu-id="b17f5-112">Wskazuje, że to polecenie cmdlet wyłącza stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b17f5-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17f5-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b17f5-113">-InformationAction</span></span>
<span data-ttu-id="b17f5-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b17f5-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b17f5-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b17f5-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b17f5-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b17f5-116">Continue</span></span>
- <span data-ttu-id="b17f5-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b17f5-117">Ignore</span></span>
- <span data-ttu-id="b17f5-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="b17f5-118">Inquire</span></span>
- <span data-ttu-id="b17f5-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b17f5-119">SilentlyContinue</span></span>
- <span data-ttu-id="b17f5-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b17f5-120">Stop</span></span>
- <span data-ttu-id="b17f5-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b17f5-121">Suspend</span></span>

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

### <span data-ttu-id="b17f5-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b17f5-122">-InformationVariable</span></span>
<span data-ttu-id="b17f5-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b17f5-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b17f5-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="b17f5-124">-Profile</span></span>
<span data-ttu-id="b17f5-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b17f5-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b17f5-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b17f5-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b17f5-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="b17f5-127">-PuppetMasterServer</span></span>
<span data-ttu-id="b17f5-128">Określa w pełni kwalifikowaną nazwę domeny (FQDN) serwera Puppet Master.</span><span class="sxs-lookup"><span data-stu-id="b17f5-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="b17f5-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b17f5-129">-ReferenceName</span></span>
<span data-ttu-id="b17f5-130">Określa nazwę referencyjną rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b17f5-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="b17f5-131">Jest to ciąg zdefiniowany przez użytkownika, który służy do odwoływania się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b17f5-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="b17f5-132">Jest ona określana po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b17f5-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="b17f5-133">W przypadku kolejnych aktualizacji należy określić poprzednio zastosowaną nazwę referencyjną podczas aktualizacji rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b17f5-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="b17f5-134">Element ReferenceName przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b17f5-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b17f5-135">-Version</span><span class="sxs-lookup"><span data-stu-id="b17f5-135">-Version</span></span>
<span data-ttu-id="b17f5-136">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="b17f5-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="b17f5-137">-VM</span><span class="sxs-lookup"><span data-stu-id="b17f5-137">-VM</span></span>
<span data-ttu-id="b17f5-138">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b17f5-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b17f5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17f5-139">CommonParameters</span></span>
<span data-ttu-id="b17f5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17f5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17f5-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b17f5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17f5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b17f5-142">INPUTS</span></span>

## <span data-ttu-id="b17f5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b17f5-143">OUTPUTS</span></span>

## <span data-ttu-id="b17f5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b17f5-144">NOTES</span></span>

## <span data-ttu-id="b17f5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b17f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="b17f5-146">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b17f5-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


