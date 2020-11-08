---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3DCA1502-9528-458D-A9EA-762A4BD2726B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284fcf4bd31eeb9437b8cc7669fff0824155180f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055414"
---
# <span data-ttu-id="3f2f0-101">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f2f0-101">Remove-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="3f2f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2f0-103">Usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-103">Removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="3f2f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f2f0-104">SYNTAX</span></span>

```
Remove-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f2f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3f2f0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f2f0-106">Polecenie cmdlet **Remove-AzureVMCustomScriptExtension** usuwa niestandardowe rozszerzenie skryptu z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-106">The **Remove-AzureVMCustomScriptExtension** cmdlet removes the custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="3f2f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f2f0-107">EXAMPLES</span></span>

### <span data-ttu-id="3f2f0-108">Przykład 1: Usuwanie niestandardowego rozszerzenia skryptu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="3f2f0-108">Example 1: Remove a virtual machine custom script extension</span></span>
```
PS C:\> Remove-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="3f2f0-109">To polecenie powoduje usunięcie niestandardowego rozszerzenia skryptu maszyny wirtualnej platformy Azure z określonej maszyny wirtualnej zapisanej w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-109">This command removes the Azure virtual machine custom script extension from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="3f2f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f2f0-110">PARAMETERS</span></span>

### <span data-ttu-id="3f2f0-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f2f0-111">-InformationAction</span></span>
<span data-ttu-id="3f2f0-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f2f0-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3f2f0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f2f0-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="3f2f0-114">Continue</span></span>
- <span data-ttu-id="3f2f0-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="3f2f0-115">Ignore</span></span>
- <span data-ttu-id="3f2f0-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="3f2f0-116">Inquire</span></span>
- <span data-ttu-id="3f2f0-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f2f0-117">SilentlyContinue</span></span>
- <span data-ttu-id="3f2f0-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="3f2f0-118">Stop</span></span>
- <span data-ttu-id="3f2f0-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="3f2f0-119">Suspend</span></span>

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

### <span data-ttu-id="3f2f0-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f2f0-120">-InformationVariable</span></span>
<span data-ttu-id="3f2f0-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f2f0-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="3f2f0-122">-Profile</span></span>
<span data-ttu-id="3f2f0-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f2f0-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f2f0-125">-VM</span><span class="sxs-lookup"><span data-stu-id="3f2f0-125">-VM</span></span>
<span data-ttu-id="3f2f0-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3f2f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2f0-127">CommonParameters</span></span>
<span data-ttu-id="3f2f0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2f0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2f0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f2f0-130">INPUTS</span></span>

## <span data-ttu-id="3f2f0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f2f0-131">OUTPUTS</span></span>

## <span data-ttu-id="3f2f0-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f2f0-132">NOTES</span></span>

## <span data-ttu-id="3f2f0-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f2f0-133">RELATED LINKS</span></span>

[<span data-ttu-id="3f2f0-134">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f2f0-134">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="3f2f0-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="3f2f0-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


