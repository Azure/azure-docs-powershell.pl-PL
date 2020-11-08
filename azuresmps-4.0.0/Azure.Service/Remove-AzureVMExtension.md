---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054467"
---
# <span data-ttu-id="9a461-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="9a461-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="9a461-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a461-102">SYNOPSIS</span></span>
<span data-ttu-id="9a461-103">Usuwa rozszerzenia zasobów z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9a461-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="9a461-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a461-104">SYNTAX</span></span>

### <span data-ttu-id="9a461-105">RemoveByExtensionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9a461-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a461-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="9a461-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9a461-107">Nad!</span><span class="sxs-lookup"><span data-stu-id="9a461-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9a461-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9a461-108">DESCRIPTION</span></span>
<span data-ttu-id="9a461-109">Polecenie cmdlet **Remove-AzureVMExtension** usuwa rozszerzenia zasobów z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9a461-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="9a461-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a461-110">EXAMPLES</span></span>

### <span data-ttu-id="9a461-111">Przykład 1: Usuwanie rozszerzenia przy użyciu określonej nazwy i wydawcy</span><span class="sxs-lookup"><span data-stu-id="9a461-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="9a461-112">To polecenie usuwa rozszerzenie o określonej nazwie i wydawcy.</span><span class="sxs-lookup"><span data-stu-id="9a461-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="9a461-113">Przykład 2: Usuwanie wszystkich rozszerzeń z określonej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9a461-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="9a461-114">To polecenie usuwa wszystkie rozszerzenia z określonej maszyny wirtualnej jako przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="9a461-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="9a461-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a461-115">PARAMETERS</span></span>

### <span data-ttu-id="9a461-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="9a461-116">-ExtensionName</span></span>
<span data-ttu-id="9a461-117">Określa nazwę rozszerzenia, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a461-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a461-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9a461-118">-InformationAction</span></span>
<span data-ttu-id="9a461-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9a461-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9a461-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9a461-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a461-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9a461-121">Continue</span></span>
- <span data-ttu-id="9a461-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9a461-122">Ignore</span></span>
- <span data-ttu-id="9a461-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="9a461-123">Inquire</span></span>
- <span data-ttu-id="9a461-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9a461-124">SilentlyContinue</span></span>
- <span data-ttu-id="9a461-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9a461-125">Stop</span></span>
- <span data-ttu-id="9a461-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9a461-126">Suspend</span></span>

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

### <span data-ttu-id="9a461-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9a461-127">-InformationVariable</span></span>
<span data-ttu-id="9a461-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9a461-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9a461-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="9a461-129">-Profile</span></span>
<span data-ttu-id="9a461-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a461-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9a461-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9a461-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9a461-132">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="9a461-132">-Publisher</span></span>
<span data-ttu-id="9a461-133">Umożliwia określenie wydawcy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9a461-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a461-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="9a461-134">-ReferenceName</span></span>
<span data-ttu-id="9a461-135">Określa nazwę referencyjną rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="9a461-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a461-136">-Wszystkie</span><span class="sxs-lookup"><span data-stu-id="9a461-136">-RemoveAll</span></span>
<span data-ttu-id="9a461-137">Wskazuje, że to polecenie cmdlet usuwa wszystkie rozszerzenia zasobów z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9a461-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a461-138">-VM</span><span class="sxs-lookup"><span data-stu-id="9a461-138">-VM</span></span>
<span data-ttu-id="9a461-139">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9a461-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="9a461-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a461-140">CommonParameters</span></span>
<span data-ttu-id="9a461-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a461-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a461-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a461-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a461-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a461-143">INPUTS</span></span>

## <span data-ttu-id="9a461-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a461-144">OUTPUTS</span></span>

## <span data-ttu-id="9a461-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a461-145">NOTES</span></span>

## <span data-ttu-id="9a461-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a461-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a461-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="9a461-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="9a461-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="9a461-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


