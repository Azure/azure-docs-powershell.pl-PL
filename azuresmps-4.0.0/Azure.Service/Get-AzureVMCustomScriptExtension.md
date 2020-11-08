---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054497"
---
# <span data-ttu-id="9e55c-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e55c-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="9e55c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e55c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e55c-103">Pobiera informacje z niestandardowego rozszerzenia skryptu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e55c-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="9e55c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e55c-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e55c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e55c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e55c-106">Polecenie cmdlet **Get-AzureVMCustomScriptExtension** pobiera informacje z niestandardowego rozszerzenia skryptu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9e55c-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="9e55c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e55c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e55c-108">Przykład 1: pobieranie rozszerzenia skryptu maszyny wirtualnej platformy Azure</span><span class="sxs-lookup"><span data-stu-id="9e55c-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="9e55c-109">To polecenie pobiera rozszerzenie skryptu maszyny wirtualnej platformy Azure przechowywane w zmiennej $VM.</span><span class="sxs-lookup"><span data-stu-id="9e55c-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="9e55c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e55c-110">PARAMETERS</span></span>

### <span data-ttu-id="9e55c-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9e55c-111">-InformationAction</span></span>
<span data-ttu-id="9e55c-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9e55c-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9e55c-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9e55c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e55c-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9e55c-114">Continue</span></span>
- <span data-ttu-id="9e55c-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9e55c-115">Ignore</span></span>
- <span data-ttu-id="9e55c-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="9e55c-116">Inquire</span></span>
- <span data-ttu-id="9e55c-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9e55c-117">SilentlyContinue</span></span>
- <span data-ttu-id="9e55c-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9e55c-118">Stop</span></span>
- <span data-ttu-id="9e55c-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9e55c-119">Suspend</span></span>

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

### <span data-ttu-id="9e55c-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9e55c-120">-InformationVariable</span></span>
<span data-ttu-id="9e55c-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9e55c-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9e55c-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="9e55c-122">-Profile</span></span>
<span data-ttu-id="9e55c-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e55c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9e55c-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9e55c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9e55c-125">-VM</span><span class="sxs-lookup"><span data-stu-id="9e55c-125">-VM</span></span>
<span data-ttu-id="9e55c-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9e55c-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="9e55c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e55c-127">CommonParameters</span></span>
<span data-ttu-id="9e55c-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e55c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e55c-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e55c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e55c-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e55c-130">INPUTS</span></span>

## <span data-ttu-id="9e55c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e55c-131">OUTPUTS</span></span>

## <span data-ttu-id="9e55c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e55c-132">NOTES</span></span>

## <span data-ttu-id="9e55c-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e55c-133">RELATED LINKS</span></span>

[<span data-ttu-id="9e55c-134">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e55c-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="9e55c-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e55c-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


