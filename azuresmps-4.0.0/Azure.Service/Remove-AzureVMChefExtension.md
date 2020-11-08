---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A46832F2-CA94-43A4-AFF9-70D02851713F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1146cee245693c19b333af5a4efd9fcc1bebc725
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054471"
---
# <span data-ttu-id="daf84-101">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="daf84-101">Remove-AzureVMChefExtension</span></span>

## <span data-ttu-id="daf84-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daf84-102">SYNOPSIS</span></span>
<span data-ttu-id="daf84-103">Usuwa rozszerzenie Kuchmistrz zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daf84-103">Removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="daf84-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daf84-104">SYNTAX</span></span>

```
Remove-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="daf84-105">Opis</span><span class="sxs-lookup"><span data-stu-id="daf84-105">DESCRIPTION</span></span>
<span data-ttu-id="daf84-106">Polecenie cmdlet **Remove-AzureVMChefExtension** usuwa rozszerzenie Kuchmistrz zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daf84-106">The **Remove-AzureVMChefExtension** cmdlet deletes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="daf84-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daf84-107">EXAMPLES</span></span>

### <span data-ttu-id="daf84-108">Przykład 1: Usuwanie rozszerzenia Kuchmistrz zastosowanego na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="daf84-108">Example 1: Remove the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Remove-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="daf84-109">To polecenie usuwa rozszerzenie Kuchmistrz zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daf84-109">This command removes the Chef extension applied on the virtual machine.</span></span>

## <span data-ttu-id="daf84-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daf84-110">PARAMETERS</span></span>

### <span data-ttu-id="daf84-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="daf84-111">-InformationAction</span></span>
<span data-ttu-id="daf84-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="daf84-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="daf84-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="daf84-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="daf84-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="daf84-114">Continue</span></span>
- <span data-ttu-id="daf84-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="daf84-115">Ignore</span></span>
- <span data-ttu-id="daf84-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="daf84-116">Inquire</span></span>
- <span data-ttu-id="daf84-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="daf84-117">SilentlyContinue</span></span>
- <span data-ttu-id="daf84-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="daf84-118">Stop</span></span>
- <span data-ttu-id="daf84-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="daf84-119">Suspend</span></span>

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

### <span data-ttu-id="daf84-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="daf84-120">-InformationVariable</span></span>
<span data-ttu-id="daf84-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="daf84-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="daf84-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="daf84-122">-Profile</span></span>
<span data-ttu-id="daf84-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf84-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="daf84-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="daf84-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="daf84-125">-VM</span><span class="sxs-lookup"><span data-stu-id="daf84-125">-VM</span></span>
<span data-ttu-id="daf84-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="daf84-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="daf84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf84-127">CommonParameters</span></span>
<span data-ttu-id="daf84-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf84-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf84-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf84-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daf84-130">INPUTS</span></span>

## <span data-ttu-id="daf84-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daf84-131">OUTPUTS</span></span>

## <span data-ttu-id="daf84-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daf84-132">NOTES</span></span>

## <span data-ttu-id="daf84-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daf84-133">RELATED LINKS</span></span>

[<span data-ttu-id="daf84-134">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="daf84-134">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="daf84-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="daf84-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


