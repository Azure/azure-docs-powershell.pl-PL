---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054562"
---
# <span data-ttu-id="f5387-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="f5387-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="f5387-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5387-102">SYNOPSIS</span></span>
<span data-ttu-id="f5387-103">To polecenie cmdlet umożliwia pobieranie rozszerzenia pulpitu zdalnego usługi w chmurze zastosowanego do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f5387-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="f5387-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5387-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f5387-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5387-105">DESCRIPTION</span></span>
<span data-ttu-id="f5387-106">Polecenie cmdlet **Get-AzureServiceRemoteDesktopExtension** pobiera rozszerzenie pulpitu zdalnego usługi w chmurze zastosowane do wszystkich ról lub nazwanych ról w określonym miejscu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f5387-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="f5387-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5387-107">EXAMPLES</span></span>

### <span data-ttu-id="f5387-108">Przykład 1: Uzyskaj rozszerzenie pulpitu zdalnego dla określonej usługi</span><span class="sxs-lookup"><span data-stu-id="f5387-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="f5387-109">To polecenie pobiera rozszerzenie pulpitu zdalnego dla określonej usługi.</span><span class="sxs-lookup"><span data-stu-id="f5387-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="f5387-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5387-110">PARAMETERS</span></span>

### <span data-ttu-id="f5387-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f5387-111">-InformationAction</span></span>
<span data-ttu-id="f5387-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="f5387-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f5387-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f5387-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5387-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="f5387-114">Continue</span></span>
- <span data-ttu-id="f5387-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="f5387-115">Ignore</span></span>
- <span data-ttu-id="f5387-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f5387-116">Inquire</span></span>
- <span data-ttu-id="f5387-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f5387-117">SilentlyContinue</span></span>
- <span data-ttu-id="f5387-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="f5387-118">Stop</span></span>
- <span data-ttu-id="f5387-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="f5387-119">Suspend</span></span>

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

### <span data-ttu-id="f5387-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f5387-120">-InformationVariable</span></span>
<span data-ttu-id="f5387-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="f5387-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f5387-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="f5387-122">-Profile</span></span>
<span data-ttu-id="f5387-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5387-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5387-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f5387-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5387-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f5387-125">-ServiceName</span></span>
<span data-ttu-id="f5387-126">Określa nazwę usługi na platformie Azure wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f5387-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="f5387-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="f5387-127">-Slot</span></span>
<span data-ttu-id="f5387-128">Określa środowisko wdrożenia, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="f5387-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="f5387-129">Dopuszczalne wartości tego parametru to: production lub Staging.</span><span class="sxs-lookup"><span data-stu-id="f5387-129">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="f5387-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5387-130">CommonParameters</span></span>
<span data-ttu-id="f5387-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5387-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5387-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5387-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5387-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5387-133">INPUTS</span></span>

## <span data-ttu-id="f5387-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5387-134">OUTPUTS</span></span>

## <span data-ttu-id="f5387-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5387-135">NOTES</span></span>

## <span data-ttu-id="f5387-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5387-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5387-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="f5387-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


