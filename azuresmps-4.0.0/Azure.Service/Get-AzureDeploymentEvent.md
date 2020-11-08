---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054616"
---
# <span data-ttu-id="48224-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="48224-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="48224-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48224-102">SYNOPSIS</span></span>
<span data-ttu-id="48224-103">Pobiera informacje na temat zdarzeń inicjowanych przez platformę Azure, które wpływają na maszyny wirtualne i usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="48224-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="48224-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48224-104">SYNTAX</span></span>

### <span data-ttu-id="48224-105">GetDeploymentEventBySlot (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48224-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="48224-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="48224-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="48224-107">Opis</span><span class="sxs-lookup"><span data-stu-id="48224-107">DESCRIPTION</span></span>
<span data-ttu-id="48224-108">Polecenie cmdlet **Get-AzureDeploymentEvent** pobiera informacje dotyczące zdarzeń inicjowanych przez platformę Azure, które wpływają na maszyny wirtualne i usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="48224-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="48224-109">Zdarzenia te obejmują zaplanowane zdarzenia konserwacji.</span><span class="sxs-lookup"><span data-stu-id="48224-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="48224-110">To polecenie cmdlet zwraca listę zdarzeń, które identyfikują dotkniętą instancję roli lub maszynę wirtualną, przyczynę wpływu oraz godzinę rozpoczęcia zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="48224-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="48224-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48224-111">EXAMPLES</span></span>

### <span data-ttu-id="48224-112">1:1</span><span class="sxs-lookup"><span data-stu-id="48224-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="48224-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48224-113">PARAMETERS</span></span>

### <span data-ttu-id="48224-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="48224-114">-DeploymentName</span></span>
<span data-ttu-id="48224-115">Określa nazwę wdrożenia, dla którego to polecenie cmdlet pobiera zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="48224-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48224-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="48224-116">-EndTime</span></span>
<span data-ttu-id="48224-117">Określa godzinę zakończenia zaplanowanego zdarzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48224-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48224-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="48224-118">-InformationAction</span></span>
<span data-ttu-id="48224-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="48224-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="48224-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="48224-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48224-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="48224-121">Continue</span></span>
- <span data-ttu-id="48224-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="48224-122">Ignore</span></span>
- <span data-ttu-id="48224-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="48224-123">Inquire</span></span>
- <span data-ttu-id="48224-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="48224-124">SilentlyContinue</span></span>
- <span data-ttu-id="48224-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="48224-125">Stop</span></span>
- <span data-ttu-id="48224-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="48224-126">Suspend</span></span>

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

### <span data-ttu-id="48224-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="48224-127">-InformationVariable</span></span>
<span data-ttu-id="48224-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="48224-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="48224-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="48224-129">-Profile</span></span>
<span data-ttu-id="48224-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48224-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48224-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="48224-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48224-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48224-132">-ServiceName</span></span>
<span data-ttu-id="48224-133">Określa nazwę usługi hostowanej, dla której to polecenie cmdlet pobiera zaplanowane zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="48224-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48224-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="48224-134">-Slot</span></span>
<span data-ttu-id="48224-135">Określa środowisko wdrożenia, dla którego to polecenie cmdlet pobiera zaplanowane zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="48224-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="48224-136">Prawidłowe wartości to: przemieszczanie i produkcja.</span><span class="sxs-lookup"><span data-stu-id="48224-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="48224-137">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="48224-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48224-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="48224-138">-StartTime</span></span>
<span data-ttu-id="48224-139">Określa godzinę rozpoczęcia zaplanowanego zdarzenia, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48224-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48224-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48224-140">CommonParameters</span></span>
<span data-ttu-id="48224-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48224-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48224-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48224-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48224-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48224-143">INPUTS</span></span>

## <span data-ttu-id="48224-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48224-144">OUTPUTS</span></span>

## <span data-ttu-id="48224-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48224-145">NOTES</span></span>

## <span data-ttu-id="48224-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48224-146">RELATED LINKS</span></span>

[<span data-ttu-id="48224-147">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="48224-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


