---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C19A1DC0-47FA-4687-B81F-315EA04AD4A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22591c1aa5a670e8f0d73f206ed6d2bcbe52c88f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054460"
---
# <span data-ttu-id="ca9b6-101">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ca9b6-101">Remove-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="ca9b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca9b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9b6-103">Usuwa rozszerzenie serwera SQL maszyny wirtualnej platformy Azure z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-103">Removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="ca9b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca9b6-104">SYNTAX</span></span>

```
Remove-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ca9b6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca9b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9b6-106">Polecenie cmdlet **Remove-AzureVMSqlServerExtension** usuwa rozszerzenie serwera SQL maszyny wirtualnej platformy Azure z obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-106">The **Remove-AzureVMSqlServerExtension** cmdlet removes an Azure virtual machine SQL Server extension from a virtual machine object.</span></span>

## <span data-ttu-id="ca9b6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca9b6-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9b6-108">1:1</span><span class="sxs-lookup"><span data-stu-id="ca9b6-108">1:</span></span>
```

```

## <span data-ttu-id="ca9b6-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca9b6-109">PARAMETERS</span></span>

### <span data-ttu-id="ca9b6-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ca9b6-110">-InformationAction</span></span>
<span data-ttu-id="ca9b6-111">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ca9b6-112">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ca9b6-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ca9b6-113">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ca9b6-113">Continue</span></span>
- <span data-ttu-id="ca9b6-114">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ca9b6-114">Ignore</span></span>
- <span data-ttu-id="ca9b6-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="ca9b6-115">Inquire</span></span>
- <span data-ttu-id="ca9b6-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ca9b6-116">SilentlyContinue</span></span>
- <span data-ttu-id="ca9b6-117">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ca9b6-117">Stop</span></span>
- <span data-ttu-id="ca9b6-118">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ca9b6-118">Suspend</span></span>

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

### <span data-ttu-id="ca9b6-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ca9b6-119">-InformationVariable</span></span>
<span data-ttu-id="ca9b6-120">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ca9b6-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ca9b6-121">-Profile</span></span>
<span data-ttu-id="ca9b6-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ca9b6-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ca9b6-124">-VM</span><span class="sxs-lookup"><span data-stu-id="ca9b6-124">-VM</span></span>
<span data-ttu-id="ca9b6-125">Określa obiekt trwałej maszyny wirtualnej, którego rozszerzenie jest usuwane.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-125">Specifies the persistent virtual machine object that this cmdlet removes the extension from.</span></span>

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

### <span data-ttu-id="ca9b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9b6-126">CommonParameters</span></span>
<span data-ttu-id="ca9b6-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9b6-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9b6-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca9b6-129">INPUTS</span></span>

## <span data-ttu-id="ca9b6-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca9b6-130">OUTPUTS</span></span>

## <span data-ttu-id="ca9b6-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca9b6-131">NOTES</span></span>

## <span data-ttu-id="ca9b6-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca9b6-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca9b6-133">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ca9b6-133">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="ca9b6-134">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ca9b6-134">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


