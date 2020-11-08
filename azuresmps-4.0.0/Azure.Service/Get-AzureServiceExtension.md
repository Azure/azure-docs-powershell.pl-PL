---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054565"
---
# <span data-ttu-id="c877b-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c877b-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="c877b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c877b-102">SYNOPSIS</span></span>
<span data-ttu-id="c877b-103">Umożliwia pobieranie rozszerzeń usługi w chmurze, które zostały zastosowane we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="c877b-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="c877b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c877b-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c877b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c877b-105">DESCRIPTION</span></span>
<span data-ttu-id="c877b-106">Polecenie cmdlet **Get-AzureServiceExtension** umożliwia pobieranie istniejących rozszerzeń usługi w chmurze, które zostaną zastosowane do wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c877b-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="c877b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c877b-107">EXAMPLES</span></span>

### <span data-ttu-id="c877b-108">Przykład 1: uzyskiwanie określonego rozszerzenia</span><span class="sxs-lookup"><span data-stu-id="c877b-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="c877b-109">To polecenie uzyskuje rozszerzenie usługi w chmurze o określonej nazwie i przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="c877b-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="c877b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c877b-110">PARAMETERS</span></span>

### <span data-ttu-id="c877b-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c877b-111">-ExtensionName</span></span>
<span data-ttu-id="c877b-112">Określa nazwę rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c877b-112">Specifies the extension name.</span></span>

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

### <span data-ttu-id="c877b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c877b-113">-InformationAction</span></span>
<span data-ttu-id="c877b-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c877b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c877b-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c877b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c877b-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c877b-116">Continue</span></span>
- <span data-ttu-id="c877b-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c877b-117">Ignore</span></span>
- <span data-ttu-id="c877b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="c877b-118">Inquire</span></span>
- <span data-ttu-id="c877b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c877b-119">SilentlyContinue</span></span>
- <span data-ttu-id="c877b-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c877b-120">Stop</span></span>
- <span data-ttu-id="c877b-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c877b-121">Suspend</span></span>

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

### <span data-ttu-id="c877b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c877b-122">-InformationVariable</span></span>
<span data-ttu-id="c877b-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c877b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c877b-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="c877b-124">-Profile</span></span>
<span data-ttu-id="c877b-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c877b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c877b-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c877b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c877b-127">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c877b-127">-ProviderNamespace</span></span>
<span data-ttu-id="c877b-128">Określa obszar nazw dostawcy rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="c877b-128">Specifies the extension provider namespace.</span></span>

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

### <span data-ttu-id="c877b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c877b-129">-ServiceName</span></span>
<span data-ttu-id="c877b-130">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c877b-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="c877b-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="c877b-131">-Slot</span></span>
<span data-ttu-id="c877b-132">Określa środowisko wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c877b-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="c877b-133">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="c877b-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="c877b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c877b-134">CommonParameters</span></span>
<span data-ttu-id="c877b-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c877b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c877b-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c877b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c877b-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c877b-137">INPUTS</span></span>

## <span data-ttu-id="c877b-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c877b-138">OUTPUTS</span></span>

## <span data-ttu-id="c877b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c877b-139">NOTES</span></span>

## <span data-ttu-id="c877b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c877b-140">RELATED LINKS</span></span>

[<span data-ttu-id="c877b-141">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c877b-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="c877b-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="c877b-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


