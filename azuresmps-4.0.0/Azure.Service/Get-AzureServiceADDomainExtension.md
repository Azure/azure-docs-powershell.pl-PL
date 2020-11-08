---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054573"
---
# <span data-ttu-id="04604-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="04604-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="04604-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04604-102">SYNOPSIS</span></span>
<span data-ttu-id="04604-103">Pobiera rozszerzenie domeny usługi Cloud Active Directory (AD), które dotyczy wszystkich ról lub ról nazwanych w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="04604-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="04604-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04604-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="04604-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04604-105">DESCRIPTION</span></span>
<span data-ttu-id="04604-106">Polecenie cmdlet **Get-AzureServiceADDomainExtension** pobiera rozszerzenie domeny usługi w chmurze, które dotyczy wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="04604-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="04604-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04604-107">EXAMPLES</span></span>

### <span data-ttu-id="04604-108">Przykład 1: uzyskiwanie rozszerzenia domeny usługi Active Directory dla określonej usługi</span><span class="sxs-lookup"><span data-stu-id="04604-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="04604-109">To polecenie uzyskuje rozszerzenie domeny usługi Active Directory dla usługi określonej w $Svc.</span><span class="sxs-lookup"><span data-stu-id="04604-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="04604-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04604-110">PARAMETERS</span></span>

### <span data-ttu-id="04604-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04604-111">-InformationAction</span></span>
<span data-ttu-id="04604-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="04604-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04604-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04604-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04604-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="04604-114">Continue</span></span>
- <span data-ttu-id="04604-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="04604-115">Ignore</span></span>
- <span data-ttu-id="04604-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="04604-116">Inquire</span></span>
- <span data-ttu-id="04604-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04604-117">SilentlyContinue</span></span>
- <span data-ttu-id="04604-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="04604-118">Stop</span></span>
- <span data-ttu-id="04604-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="04604-119">Suspend</span></span>

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

### <span data-ttu-id="04604-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04604-120">-InformationVariable</span></span>
<span data-ttu-id="04604-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="04604-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="04604-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="04604-122">-Profile</span></span>
<span data-ttu-id="04604-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04604-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04604-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="04604-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04604-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="04604-125">-ServiceName</span></span>
<span data-ttu-id="04604-126">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="04604-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04604-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="04604-127">-Slot</span></span>
<span data-ttu-id="04604-128">Określa środowisko wdrażania.</span><span class="sxs-lookup"><span data-stu-id="04604-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="04604-129">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="04604-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04604-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04604-130">CommonParameters</span></span>
<span data-ttu-id="04604-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04604-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04604-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04604-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04604-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04604-133">INPUTS</span></span>

## <span data-ttu-id="04604-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04604-134">OUTPUTS</span></span>

## <span data-ttu-id="04604-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04604-135">NOTES</span></span>

## <span data-ttu-id="04604-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04604-136">RELATED LINKS</span></span>

[<span data-ttu-id="04604-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="04604-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="04604-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="04604-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


