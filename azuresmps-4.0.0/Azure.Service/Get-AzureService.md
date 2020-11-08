---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055275"
---
# <span data-ttu-id="39810-101">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="39810-101">Get-AzureService</span></span>

## <span data-ttu-id="39810-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39810-102">SYNOPSIS</span></span>
<span data-ttu-id="39810-103">Zwraca obiekt z informacją o usługach w chmurze dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="39810-103">Returns an object with information about the cloud services for the current subscription.</span></span>

## <span data-ttu-id="39810-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39810-104">SYNTAX</span></span>

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="39810-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39810-105">DESCRIPTION</span></span>
<span data-ttu-id="39810-106">Polecenie cmdlet **Get-AzureService** zwraca obiekt listy ze wszystkimi usługami usługi Azure Cloud skojarzonymi z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="39810-106">The **Get-AzureService** cmdlet returns a list object with all of the Azure cloud services associated with the current subscription.</span></span>
<span data-ttu-id="39810-107">Jeśli określisz parametr *ServiceName* , funkcja **Get-AzureService** zwraca informacje dotyczące tylko usługi zgodnej.</span><span class="sxs-lookup"><span data-stu-id="39810-107">If you specify the *ServiceName* parameter, **Get-AzureService** returns information on only the matching service.</span></span>

## <span data-ttu-id="39810-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39810-108">EXAMPLES</span></span>

### <span data-ttu-id="39810-109">Przykład 1: uzyskiwanie informacji o wszystkich usługach</span><span class="sxs-lookup"><span data-stu-id="39810-109">Example 1: Get information about all services</span></span>
```
PS C:\> Get-AzureService
```

<span data-ttu-id="39810-110">To polecenie zwraca obiekt zawierający informacje dotyczące wszystkich usług platformy Azure skojarzonych z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="39810-110">This command returns an object that contains information about all of the Azure services associated with the current subscription.</span></span>

### <span data-ttu-id="39810-111">Przykład 2: uzyskiwanie informacji o określonej usłudze</span><span class="sxs-lookup"><span data-stu-id="39810-111">Example 2: Get information about a specified service</span></span>
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

<span data-ttu-id="39810-112">To polecenie zwraca informacje o usłudze $MySvc.</span><span class="sxs-lookup"><span data-stu-id="39810-112">This command returns information about the $MySvc service.</span></span>

### <span data-ttu-id="39810-113">Przykład 3: wyświetlanie dostępnych metod i właściwości</span><span class="sxs-lookup"><span data-stu-id="39810-113">Example 3: Display available methods and properties</span></span>
```
PS C:\> Get-AzureService | Get-Member
```

<span data-ttu-id="39810-114">To polecenie wyświetla właściwości i metody dostępne w polecenia cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="39810-114">This command displays the properties and methods that are available from the **Get-AzureService** cmdlet.</span></span>

## <span data-ttu-id="39810-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39810-115">PARAMETERS</span></span>

### <span data-ttu-id="39810-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="39810-116">-InformationAction</span></span>
<span data-ttu-id="39810-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="39810-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="39810-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="39810-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39810-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="39810-119">Continue</span></span>
- <span data-ttu-id="39810-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="39810-120">Ignore</span></span>
- <span data-ttu-id="39810-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="39810-121">Inquire</span></span>
- <span data-ttu-id="39810-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="39810-122">SilentlyContinue</span></span>
- <span data-ttu-id="39810-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="39810-123">Stop</span></span>
- <span data-ttu-id="39810-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="39810-124">Suspend</span></span>

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

### <span data-ttu-id="39810-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="39810-125">-InformationVariable</span></span>
<span data-ttu-id="39810-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="39810-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="39810-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="39810-127">-Profile</span></span>
<span data-ttu-id="39810-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39810-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39810-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="39810-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39810-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="39810-130">-ServiceName</span></span>
<span data-ttu-id="39810-131">Określa nazwę usługi, na której należy zwrócić informacje.</span><span class="sxs-lookup"><span data-stu-id="39810-131">Specifies the name of a service on which to return information.</span></span>

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

### <span data-ttu-id="39810-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39810-132">CommonParameters</span></span>
<span data-ttu-id="39810-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39810-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39810-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39810-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39810-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39810-135">INPUTS</span></span>

## <span data-ttu-id="39810-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39810-136">OUTPUTS</span></span>

### <span data-ttu-id="39810-137">HostedServiceContext</span><span class="sxs-lookup"><span data-stu-id="39810-137">HostedServiceContext</span></span>

## <span data-ttu-id="39810-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39810-138">NOTES</span></span>

## <span data-ttu-id="39810-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39810-139">RELATED LINKS</span></span>

[<span data-ttu-id="39810-140">Nowe — AzureService</span><span class="sxs-lookup"><span data-stu-id="39810-140">New-AzureService</span></span>](./New-AzureService.md)

[<span data-ttu-id="39810-141">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="39810-141">Set-AzureService</span></span>](./Set-AzureService.md)


