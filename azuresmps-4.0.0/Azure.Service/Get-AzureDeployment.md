---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055321"
---
# <span data-ttu-id="a79f2-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a79f2-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="a79f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a79f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a79f2-103">Pobiera szczegóły wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a79f2-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="a79f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a79f2-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a79f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a79f2-105">DESCRIPTION</span></span>
<span data-ttu-id="a79f2-106">Polecenie cmdlet **Get-AzureDeployment** pobiera szczegółowe informacje o wdrożeniu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a79f2-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="a79f2-107">Określ nazwę usługi Azure oraz miejsce wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a79f2-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="a79f2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a79f2-108">EXAMPLES</span></span>

### <span data-ttu-id="a79f2-109">Przykład 1: uzyskiwanie szczegółowych informacji o wdrożeniu produkcji</span><span class="sxs-lookup"><span data-stu-id="a79f2-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="a79f2-110">To polecenie zwraca szczegóły wdrożenia usługi o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="a79f2-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="a79f2-111">To polecenie nie określa gniazda.</span><span class="sxs-lookup"><span data-stu-id="a79f2-111">This command does not specify a slot.</span></span>
<span data-ttu-id="a79f2-112">Dlatego w poleceniu użyto wartości domyślnej produkcja.</span><span class="sxs-lookup"><span data-stu-id="a79f2-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="a79f2-113">Przykład 2: uzyskiwanie szczegółowych informacji dotyczących wdrożenia przemieszczania</span><span class="sxs-lookup"><span data-stu-id="a79f2-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="a79f2-114">To polecenie zwraca szczegóły przemieszczania wdrożenia ContosoService.</span><span class="sxs-lookup"><span data-stu-id="a79f2-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="a79f2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a79f2-115">PARAMETERS</span></span>

### <span data-ttu-id="a79f2-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a79f2-116">-InformationAction</span></span>
<span data-ttu-id="a79f2-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a79f2-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a79f2-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a79f2-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a79f2-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a79f2-119">Continue</span></span>
- <span data-ttu-id="a79f2-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a79f2-120">Ignore</span></span>
- <span data-ttu-id="a79f2-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="a79f2-121">Inquire</span></span>
- <span data-ttu-id="a79f2-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a79f2-122">SilentlyContinue</span></span>
- <span data-ttu-id="a79f2-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a79f2-123">Stop</span></span>
- <span data-ttu-id="a79f2-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a79f2-124">Suspend</span></span>

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

### <span data-ttu-id="a79f2-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a79f2-125">-InformationVariable</span></span>
<span data-ttu-id="a79f2-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a79f2-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a79f2-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="a79f2-127">-Profile</span></span>
<span data-ttu-id="a79f2-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a79f2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a79f2-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a79f2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a79f2-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a79f2-130">-ServiceName</span></span>
<span data-ttu-id="a79f2-131">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="a79f2-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="a79f2-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="a79f2-132">-Slot</span></span>
<span data-ttu-id="a79f2-133">Określa środowisko wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a79f2-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="a79f2-134">Prawidłowe wartości to: przemieszczanie lub produkcja.</span><span class="sxs-lookup"><span data-stu-id="a79f2-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="a79f2-135">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="a79f2-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79f2-136">CommonParameters</span></span>
<span data-ttu-id="a79f2-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79f2-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a79f2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79f2-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a79f2-139">INPUTS</span></span>

## <span data-ttu-id="a79f2-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a79f2-140">OUTPUTS</span></span>

## <span data-ttu-id="a79f2-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a79f2-141">NOTES</span></span>

## <span data-ttu-id="a79f2-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a79f2-142">RELATED LINKS</span></span>

[<span data-ttu-id="a79f2-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="a79f2-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="a79f2-144">Przenieś — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a79f2-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="a79f2-145">Nowe — AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a79f2-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="a79f2-146">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a79f2-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="a79f2-147">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="a79f2-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


