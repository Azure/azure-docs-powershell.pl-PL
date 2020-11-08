---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1721107D-22FF-4A42-93C6-FD812DF81C33
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac1bb63645b8db9e6a66971ad4ecd3b545a39100
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055511"
---
# <span data-ttu-id="350fc-101">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="350fc-101">Get-AzureVMChefExtension</span></span>

## <span data-ttu-id="350fc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="350fc-102">SYNOPSIS</span></span>
<span data-ttu-id="350fc-103">Pobiera rozszerzenie Kuchmistrz zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="350fc-103">Gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="350fc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="350fc-104">SYNTAX</span></span>

```
Get-AzureVMChefExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="350fc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="350fc-105">DESCRIPTION</span></span>
<span data-ttu-id="350fc-106">Polecenie cmdlet **Get-AzureVMChefExtension** pobiera rozszerzenie Kuchmistrz zastosowane na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="350fc-106">The **Get-AzureVMChefExtension** cmdlet gets the Chef extension applied on a virtual machine.</span></span>

## <span data-ttu-id="350fc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="350fc-107">EXAMPLES</span></span>

### <span data-ttu-id="350fc-108">Przykład 1: uzyskiwanie rozszerzenia Kuchmistrz zastosowanego na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="350fc-108">Example 1: Get the Chef extension applied on the specified virtual machine</span></span>
```
PS C:\> Get-AzureVMChefExtension -VM $VM;
```

<span data-ttu-id="350fc-109">To polecenie pobiera rozszerzenie Kuchmistrz zastosowane na określonej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="350fc-109">This command gets the Chef extension applied on the specified virtual machine.</span></span>

## <span data-ttu-id="350fc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="350fc-110">PARAMETERS</span></span>

### <span data-ttu-id="350fc-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="350fc-111">-InformationAction</span></span>
<span data-ttu-id="350fc-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="350fc-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="350fc-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="350fc-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="350fc-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="350fc-114">Continue</span></span>
- <span data-ttu-id="350fc-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="350fc-115">Ignore</span></span>
- <span data-ttu-id="350fc-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="350fc-116">Inquire</span></span>
- <span data-ttu-id="350fc-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="350fc-117">SilentlyContinue</span></span>
- <span data-ttu-id="350fc-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="350fc-118">Stop</span></span>
- <span data-ttu-id="350fc-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="350fc-119">Suspend</span></span>

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

### <span data-ttu-id="350fc-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="350fc-120">-InformationVariable</span></span>
<span data-ttu-id="350fc-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="350fc-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="350fc-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="350fc-122">-Profile</span></span>
<span data-ttu-id="350fc-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="350fc-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="350fc-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="350fc-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="350fc-125">-VM</span><span class="sxs-lookup"><span data-stu-id="350fc-125">-VM</span></span>
<span data-ttu-id="350fc-126">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="350fc-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="350fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="350fc-127">CommonParameters</span></span>
<span data-ttu-id="350fc-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="350fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="350fc-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="350fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="350fc-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="350fc-130">INPUTS</span></span>

## <span data-ttu-id="350fc-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="350fc-131">OUTPUTS</span></span>

## <span data-ttu-id="350fc-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="350fc-132">NOTES</span></span>

## <span data-ttu-id="350fc-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="350fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="350fc-134">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="350fc-134">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)

[<span data-ttu-id="350fc-135">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="350fc-135">Set-AzureVMChefExtension</span></span>](./Set-AzureVMChefExtension.md)


